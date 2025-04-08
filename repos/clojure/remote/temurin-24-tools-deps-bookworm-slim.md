## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:5c5f29669314ba3315c655b5f6778282f59f1cb454c48b9f28ca9661b87ac7da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fd9a5aa329b6272dd30aba140aec76211e33f9e3ee9df3d03e94a2494787dc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187705682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955537d29b471453b3d2becd1ff5934cd747863fb3722cedb3e64589714be3bd`
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0be7d4ba871b58c198a66ea044a3318771397121f69ae6bde737ec81f9b150`  
		Last Modified: Tue, 08 Apr 2025 01:36:59 GMT  
		Size: 89.9 MB (89949035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17b24f15db2b1d4b29f27a4138ca73d13b92ef6e903d74f10e60e27d74a2a6a`  
		Last Modified: Tue, 08 Apr 2025 01:36:59 GMT  
		Size: 69.5 MB (69528347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea6d4862de01f97c3644c5da906a86159d7b8074ecf6074e91c1495156d5179`  
		Last Modified: Tue, 08 Apr 2025 01:36:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28323bd7b90685f9daf90a23e4fcc0435d19aeba1bfa24ea86d52edd9915ef66`  
		Last Modified: Tue, 08 Apr 2025 01:36:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8eca95e8fc5268f6713dcbfc209644077d86d56310db8231085e390e34952933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083dd07ccff7e36ebf45f37e35b81ae2cf479e31350092ffb1d8a80d4bf90d1e`

```dockerfile
```

-	Layers:
	-	`sha256:1630b018da9cf67288d5e8547f6f1aba9cdc9bbfa01ca1423c6d620deccfea99`  
		Last Modified: Tue, 08 Apr 2025 01:36:57 GMT  
		Size: 4.9 MB (4864597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61369e04e7eb8aa9fbb2a717f1c4a01ab0fbdb634a6884e34c57113a3f7e1bb4`  
		Last Modified: Tue, 08 Apr 2025 01:36:56 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:40040e733821c2b256ad5ef2af5f1380d1acf5561e9c62eb7423ac4d7e86f3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186537959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6065f68a17cc4752653e6e56f965a88cd78f2fdb3788496da453fd80170090ad`
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e18d2baa19d8ecbec452c63857469775a49da49a6ee666e57c904c334e09651`  
		Last Modified: Tue, 08 Apr 2025 11:37:59 GMT  
		Size: 89.1 MB (89092706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8b72610d2e24e47ea16af34788db18c5f97f49058558de1c29ee337e209be1`  
		Last Modified: Tue, 08 Apr 2025 11:41:00 GMT  
		Size: 69.4 MB (69377892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a07018a3c75cbf8ea9f5cfd09ba3fea6edb6b5118709b1e295bbb8229a4f22`  
		Last Modified: Tue, 08 Apr 2025 11:40:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95eb54552fa92d97cc71cfa2f7299852941f06e387988b412875ef3e0fab6cb`  
		Last Modified: Tue, 08 Apr 2025 11:40:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c138311dfa9d48bad946d9ad48526fd1040c9b57354439d560e74b26c5e6911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314b34c555019f89dbce7c66b51d38cf384d8219f66562ae62615ed371cd676`

```dockerfile
```

-	Layers:
	-	`sha256:4b53d5a1cf6d1c9f10cdafc33e97a1d2af8eedacc0174513f63569a15fc2f82e`  
		Last Modified: Tue, 08 Apr 2025 11:40:58 GMT  
		Size: 4.9 MB (4870355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:444cafef7da568f8a6a77469d4c7b32774a68a6726a2aa3f45e8c77e2fb77826`  
		Last Modified: Tue, 08 Apr 2025 11:40:58 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
