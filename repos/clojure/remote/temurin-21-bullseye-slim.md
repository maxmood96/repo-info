## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:2078e21481255f19c40616ed277341ad4739900cafab9a35abbed7057df231cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:18df9347fc3b2cbca89a5765717dc1e93189af28b80334c662ffe5c745f09bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247299940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888b347ac069cb63036398ac84897574cdcf28a0d65dfa0e82b42a6a1e03ba54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:36:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:00 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:13 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55d10714d77b1873d00a2adf93ca24209ba44ebe16f8e9ae57e36f03912ba71`  
		Last Modified: Mon, 09 Mar 2026 20:36:37 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33137236b6c7f4c3791899c1698948e32637c633e0beb200ea9efd809f218c4d`  
		Last Modified: Mon, 09 Mar 2026 20:36:34 GMT  
		Size: 59.2 MB (59183435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5864fbe9c2759a453c0b0ddee32b83d737126c95d8cd6972394626b36d40cfd3`  
		Last Modified: Mon, 09 Mar 2026 20:36:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e6e7a300a09a52ba8def53a30bcd6e026a3d778f8740da9732b3b5a2bcfff2`  
		Last Modified: Mon, 09 Mar 2026 20:36:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46a9678c1f0053509d752846b59ccf02d443f22017c639735eece7f03d96ddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c6ef3a8fb543f564da553f2429bc2bc1901e9a56433aa6a84aeab834cc9cbe`

```dockerfile
```

-	Layers:
	-	`sha256:d594dc7d92047029070e121e86d3e5b52390f0122733a13b2ea85863f9d03f89`  
		Last Modified: Mon, 09 Mar 2026 20:36:31 GMT  
		Size: 5.3 MB (5323529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7ddb5928a7f2afc200563c0d534d0bcae8c6905e2f06dc37843d73ea0fde7c`  
		Last Modified: Mon, 09 Mar 2026 20:36:31 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2a72801ec53f927b28e2707f35815b6b35068acc25174afdbc76a0a68fc86d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244202208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3a7c1cee67bc30059b2173bfd26a0f409df330f10fa6f8f0e00518a631557d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 09 Mar 2026 20:35:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:53 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:07 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267dc3324579de6eb49a76ecbc655a214ddd25bcd9025d6442f21ce90a334c90`  
		Last Modified: Mon, 09 Mar 2026 20:36:29 GMT  
		Size: 156.1 MB (156133017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a29adb26cc5fa32a7add8423a35fc7f09afe6136bac70b5d164aa1425044f8b`  
		Last Modified: Mon, 09 Mar 2026 20:36:28 GMT  
		Size: 59.3 MB (59323678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3f141e973f49b7e5c791bfdbbce42294aa739627ac2298a5ab8262c9e1202d`  
		Last Modified: Mon, 09 Mar 2026 20:36:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b54eef2b925712f1618994ebe001ad17a6d51bce23940092f9f277ab22817e`  
		Last Modified: Mon, 09 Mar 2026 20:36:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e45fb75af1dfd736f8a150dbbe21c189a55581dea5e86a15a9f694e5693ca315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5345215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0beaabd1c2cd8f9c7c46598bee1d42fe32eb83c8436e962c72f8337a017526`

```dockerfile
```

-	Layers:
	-	`sha256:92acf80dc0e7b2ca81ec35eb7fe2bbe6379cf79a547981229e62d12053c0fa0f`  
		Last Modified: Mon, 09 Mar 2026 20:36:25 GMT  
		Size: 5.3 MB (5329261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b37530ecb37cbb5017c9cdfb4cfa0edfa23485b56a594936c9e27280d3b237f`  
		Last Modified: Mon, 09 Mar 2026 20:36:25 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
