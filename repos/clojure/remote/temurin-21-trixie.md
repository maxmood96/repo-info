## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:265bc25ffecbfecb9044d93c562fd194f63043524b695ef0fa6c09c7c6c2e061
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4a1d307fdaf6ff387c2bec11c3cc83c55aeac519141a8daea9097ae4554975fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292143989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2bcb5e4c87f8b652d90e7a6299526c35b164e0ed6b0b75c14f4f12886323644`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Mon, 28 Apr 2025 21:08:35 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c29560bcb0a94f49db0b99cdf4839c10a64961f9b16f2d4da6cf47de1a3cc5`  
		Last Modified: Tue, 13 May 2025 17:54:05 GMT  
		Size: 157.6 MB (157634543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e987d0d7bfd2d027f00d685bd1f7b713bb3f46c000763dea9a3b6e61983552ed`  
		Last Modified: Tue, 13 May 2025 17:54:04 GMT  
		Size: 85.3 MB (85260165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57ecda5f595b7e4fea0f906d21b1074c9392989f9b3c9ca858c1991477d4b15`  
		Last Modified: Tue, 13 May 2025 17:54:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3d0270decc297afb1ae61c57ebe9bae094988a9caf65404e2bcaa0527a1561`  
		Last Modified: Tue, 13 May 2025 17:54:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:efaa00caaa71c0c34b3db6cf5ab2a84a53aa890910043b36ca939306c4ffb4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7289404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0561011948e806b36f8ca7796e780b8fe0845a300cf574901ae48b2c3fb4725c`

```dockerfile
```

-	Layers:
	-	`sha256:73a73f2a989c254d55bf990e91768ef9295f7b8d646bcbce3ce8dfbc5b81d8f0`  
		Last Modified: Tue, 13 May 2025 17:54:02 GMT  
		Size: 7.3 MB (7272939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af540f704c3f86cfae28faf901a0ff5848c3a2576a4385b01c1710f18fc68a1e`  
		Last Modified: Tue, 13 May 2025 17:54:02 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af12fbb841e51b97c5dbae42a999457484829eb5ade8fd3547c9693658bd8737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290726422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b02d5e8bc5806c52d8cc468a7f05d82f93e64f750496e2c01c7e7eae3616bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676c3e417baafaf8b730adc6d0f78dc3fa5bdbb2f54632cf85169f85047e3825`  
		Last Modified: Tue, 13 May 2025 18:04:24 GMT  
		Size: 155.9 MB (155928808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1a01c6ad14d6ff0ffa6af0dc5d67dddc139e939d67b6e2723672993ab8debe`  
		Last Modified: Tue, 13 May 2025 18:06:37 GMT  
		Size: 85.2 MB (85172457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f9716b24e7995becaf5b62afd017d09ac2c1ed1ce9599acab5cd405cdc6b88`  
		Last Modified: Tue, 13 May 2025 18:06:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769dd8d09e972edacf7d5e6219f401b4ff4aa0ce935d1fbea7e00886cbfe7cc`  
		Last Modified: Tue, 13 May 2025 18:06:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:26fa8e7b45ace23d6e48b2e93fcdec2c550fefad929b6368a7165ba263dc053a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7296600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b311074def9ebbd6bd231d961cac5da839534ae84799fcffd75025f5d3667e16`

```dockerfile
```

-	Layers:
	-	`sha256:6552a24acd51053818384e1a34d1100ad89af33906624b6f068242659ec6b337`  
		Last Modified: Tue, 13 May 2025 18:06:35 GMT  
		Size: 7.3 MB (7279993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0304755cf1ff133a54a6bea45ab41a2da880ac70dce8e8552e0167da932a67`  
		Last Modified: Tue, 13 May 2025 18:06:34 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json
